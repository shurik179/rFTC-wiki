# Continuous Motion Servos
*go back to [/r/FTC wiki](/r/FTC/wiki)*

__This article is up to date as of Dec 1, 2017.__

Continuous Rotation (CR) servos are incredibly useful when you need motor-like movement but don't have the room for a full motor. For this reason we found ourselves using them a lot in our robot for everything from ball intake to beacon pokers. In order to get them to work we often had to correct misalignment in the physical servo with code. Here is how we did it. 

#### How Servos and CR Servos work
Servos are a small motor, that through a potentiometer, has it's range limited. The potentiometer turns as the motor does; thus, once the motor reaches the min or max distance, the potientiometer's resistance changes. This then tells the control circuit to stop power to the motor. A CR Servo is a servo that has had it's potentiometer removed or broken, so the control circuit always believes that the motor is at it's central position. Thus, the motor will continue to spin, resulting in the CR Servo

#### Correcting Misaligned CR Servos
Some CR servos, when they recieve the value that normally would result in them stopping, instead continue to turn. This is the result of an incorrectly calibrated potentiometer/control circuit. To fix this, a slight offset for the center value must be used. For example, using the code `crservo.setPower(0)` will not result in the motor stopping. Instead, something like `crservo.setPower(-.01)` or `crservo.setPower(.01)` will. This is one way to make the CR Servo stop. 
Another method is to declare a CR Servo as a regular servo, as in `private Servo crservo`. Hardware wise, there is a CR Servo, but you use the servo methods in the code. Since a CR Servo is just a Servo that always thinks it's the center, the servo methods can be used to control it as well. `crservo.setPosition(.5)` would stop it, in theory. However, this may not be correct. To correct this, a value near .5 may have to be used. One CR Servo had `crservo.setPosition(.48)` as the code to seize movement. To make it move, use a position skewed to one side of the center value. The farther away the position is to the center value, the faster the movement of the CR Servo. The easiest way to find this value is to create a TeleOp with two buttons to raise and lower a variable, then set the CR Servo's position to that variable. An implementation of this can be found at the bottom of the page.

***

    package org.firstinspires.ftc.teamcode;

    import com.qualcomm.robotcore.eventloop.opmode.Disabled;
    import com.qualcomm.robotcore.eventloop.opmode.OpMode;
    import com.qualcomm.robotcore.eventloop.opmode.TeleOp;
    import com.qualcomm.robotcore.hardware.Servo;
    import com.qualcomm.robotcore.util.ElapsedTime;

    @TeleOp(name="Telebop_ServoAlign", group="TESTING")
    //Note if you are using this make sure to comment out the @Disabled below or it won't show up on your phone.
    @Disabled
    public class Testing_ServoAlign extends OpMode 
    {
        //Declare a servo to represent your CRServo
        private Servo ourCrServo = null;

        //Used to add a cooldown to the button, so it won't trigger so quickly
        //Thus you can actually finely control the values
        private long pressTracker = 0;

        //The position the Cr servo will be set to
        private double position = .5;
        @Override
        public void init()
        {
            telemetry.addData("Status", "Initialized");
            // The name of the crservo in the robot config on your robot controller phone
            // Note: despite being a crservo we still choose "servo" from the dropdown in the phone

            ourCrServo = hardwareMap.servo.get("our servo");
        }


        @Override
        public void init_loop() {}

        @Override
        public void start() {}

        @Override
        public void loop() {
            //We check if the time since the last button press is greater than 500 ms, and that the button is down
            if (gamepad1.dpad_down && System.currentTimeMillis() - pressTracker > 500) {
            //Reset last button press time
            pressTracker = System.currentTimeMillis();

            //Decrement position, since dpad_down
            position = position - .01;
        } else if (gamepad1.dpad_up && System.currentTimeMillis() - pressTracker > 500) {
            //Reset last button press time
            pressTracker = System.currentTimeMillis();

            //Increment position, since dpad_up
            position = position + .01;
        }

            ourCrServo.setPosition(position);

            //The current value of position to telemetry
            telemetry.addData("Current Position", position);
            telemetry.update();
        }

        @Override
        public void stop() {}
    }


*All content on this wiki is licensed under the [Creative Commons Attribution-ShareAlike 4.0](https://creativecommons.org/licenses/by-sa/4.0/) liscense.*
/r/FTC thanks you for reading this article and asks you to [contribute](https://github.com/GeekyStudios/rFTC-wiki) soon.
