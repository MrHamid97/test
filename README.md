# Pyrogram docs:

docs.kurigram.live
copy_message() - Kurigram
3 - 4 minutes

Toggle table of contents sidebar

Client.copy_message()¶

    Copy messages of any kind.

    The method is analogous to the method forward_messages(), but the copied message doesn’t have a link to the original message.
    Usable by Users Bots

    Parameters:

            chat_id (int | str) – Unique identifier (int) or username (str) of the target chat. For your personal cloud (Saved Messages) you can simply use “me” or “self”. For a contact that exists in your Telegram address book you can use his phone number (str).

            from_chat_id (int | str) – Unique identifier (int) or username (str) of the source chat where the original message was sent. For your personal cloud (Saved Messages) you can simply use “me” or “self”. For a contact that exists in your Telegram address book you can use his phone number (str).

            message_id (int) – Message identifier in the chat specified in from_chat_id.

            caption (string, optional) – New caption for media, 0-1024 characters after entities parsing. If not specified, the original caption is kept. Pass “” (empty string) to remove the caption.

            parse_mode (ParseMode, optional) – By default, texts are parsed using both Markdown and HTML styles. You can combine both syntaxes together.

            caption_entities (List of MessageEntity) – List of special entities that appear in the new caption, which can be specified instead of parse_mode.

            disable_notification (bool, optional) – Sends the message silently. Users will receive a notification with no sound.

            message_thread_id (int, optional) – Unique identifier for the target message thread (topic) of the forum. For supergroups only.

            reply_to_message_id (int, optional) – If the message is a reply, ID of the original message.

            reply_to_chat_id (int, optional) – If the message is a reply, ID of the original chat.

            schedule_date (datetime, optional) – Date when the message will be automatically sent.

            protect_content (bool, optional) – Protects the contents of the sent message from forwarding and saving.

            has_spoiler (bool, optional) – True, if the message media is covered by a spoiler animation.

            show_caption_above_media (bool, optional) – If True, caption must be shown above the message media.

            business_connection_id (str, optional) – Unique identifier of the business connection on behalf of which the message will be sent.

            reply_markup (InlineKeyboardMarkup | ReplyKeyboardMarkup | ReplyKeyboardRemove | ForceReply, optional) – Additional interface options. An object for an inline keyboard, custom reply keyboard, instructions to remove reply keyboard or to force a reply from the user.

            allow_paid_broadcast (bool, optional) – If True, you will be allowed to send up to 1000 messages per second. Ignoring broadcasting limits for a fee of 0.1 Telegram Stars per message. The relevant Stars will be withdrawn from the bot’s balance. For bots only.

            paid_message_star_count (int, optional) – The number of Telegram Stars the user agreed to pay to send the messages.

    Returns:

        Message – On success, the copied message is returned.

    Example

    # Copy a message
    await app.copy_message(to_chat, from_chat, 123)


docs.kurigram.live
copy_media_group() - Kurigram
3 minutes

Toggle table of contents sidebar

Client.copy_media_group()¶

    Copy a media group by providing one of the message ids.
    Usable by Users Bots

    Parameters:

            chat_id (int | str) – Unique identifier (int) or username (str) of the target chat. For your personal cloud (Saved Messages) you can simply use “me” or “self”. For a contact that exists in your Telegram address book you can use his phone number (str).

            from_chat_id (int | str) – Unique identifier (int) or username (str) of the source chat where the original media group was sent. For your personal cloud (Saved Messages) you can simply use “me” or “self”. For a contact that exists in your Telegram address book you can use his phone number (str).

            message_id (int) – Message identifier in the chat specified in from_chat_id.

            captions (str | List of str , optional) – New caption for media, 0-1024 characters after entities parsing for each media. If not specified, the original caption is kept. Pass “” (empty string) to remove the caption.

            If a string is passed, it becomes a caption only for the first media. If a list of string passed, each element becomes caption for each media element. You can pass None in list to keep the original caption (see examples below).

            disable_notification (bool, optional) – Sends the message silently. Users will receive a notification with no sound.

            message_thread_id (int, optional) – Unique identifier for the target message thread (topic) of the forum. For supergroups only.

            reply_parameters (ReplyParameters, optional) – Describes reply parameters for the message that is being sent.

            schedule_date (datetime, optional) – Date when the message will be automatically sent.

            show_caption_above_media (bool, optional) – Pass True, if the caption must be shown above the message media.

            allow_paid_broadcast (bool, optional) – If True, you will be allowed to send up to 1000 messages per second. Ignoring broadcasting limits for a fee of 0.1 Telegram Stars per message. The relevant Stars will be withdrawn from the bot’s balance. For bots only.

            paid_message_star_count (int, optional) – The number of Telegram Stars the user agreed to pay to send the messages.

    Returns:

        List of Message – On success, a list of copied messages is returned.

    Example

    # Copy a media group
    await app.copy_media_group(to_chat, from_chat, 123)

    await app.copy_media_group(to_chat, from_chat, 123, captions="single caption")

    await app.copy_media_group(to_chat, from_chat, 123,
        captions=["caption 1", None, ""])



docs.kurigram.live
send_photo() - Kurigram
5 - 6 minutes

Toggle table of contents sidebar

Client.send_photo()¶

    Send photos.
    Usable by Users Bots

    Parameters:

            chat_id (int | str) – Unique identifier (int) or username (str) of the target chat. For your personal cloud (Saved Messages) you can simply use “me” or “self”. For a contact that exists in your Telegram address book you can use his phone number (str).

            photo (str | BinaryIO) – Photo to send. Pass a file_id as string to send a photo that exists on the Telegram servers, pass an HTTP URL as a string for Telegram to get a photo from the Internet, pass a file path as string to upload a new photo that exists on your local machine, or pass a binary file-like object with its attribute “.name” set for in-memory uploads.

            caption (str, optional) – Photo caption, 0-1024 characters.

            parse_mode (ParseMode, optional) – By default, texts are parsed using both Markdown and HTML styles. You can combine both syntaxes together.

            caption_entities (List of MessageEntity) – List of special entities that appear in the caption, which can be specified instead of parse_mode.

            has_spoiler (bool, optional) – Pass True if the photo needs to be covered with a spoiler animation.

            ttl_seconds (int, optional) – Self-Destruct Timer. If you set a timer, the photo will self-destruct in ttl_seconds seconds after it was viewed.

            disable_notification (bool, optional) – Sends the message silently. Users will receive a notification with no sound.

            message_thread_id (int, optional) – Unique identifier for the target message thread (topic) of the forum. For forums only.

            direct_messages_topic_id (int, optional) – Unique identifier of the topic in a channel direct messages chat administered by the current user. For directs only only.

            effect_id (int, optional) – Unique identifier of the message effect. For private chats only.

            show_caption_above_media (bool, optional) – Pass True, if the caption must be shown above the message media.

            reply_parameters (ReplyParameters, optional) – Describes reply parameters for the message that is being sent.

            schedule_date (datetime, optional) – Date when the message will be automatically sent.

            protect_content (bool, optional) – Protects the contents of the sent message from forwarding and saving.

            view_once (bool, optional) – Self-Destruct Timer. If True, the photo will self-destruct after it was viewed.

            business_connection_id (str, optional) – Unique identifier of the business connection on behalf of which the message will be sent.

            allow_paid_broadcast (bool, optional) – If True, you will be allowed to send up to 1000 messages per second. Ignoring broadcasting limits for a fee of 0.1 Telegram Stars per message. The relevant Stars will be withdrawn from the bot’s balance. For bots only.

            paid_message_star_count (int, optional) – The number of Telegram Stars the user agreed to pay to send the messages.

            suggested_post_parameters (SuggestedPostParameters, optional) – Information about the suggested post.

            reply_markup (InlineKeyboardMarkup | ReplyKeyboardMarkup | ReplyKeyboardRemove | ForceReply, optional) – Additional interface options. An object for an inline keyboard, custom reply keyboard, instructions to remove reply keyboard or to force a reply from the user.

            progress (Callable, optional) – Pass a callback function to view the file transmission progress. The function must take (current, total) as positional arguments (look at Other Parameters below for a detailed description) and will be called back each time a new file chunk has been successfully transmitted.

            progress_args (tuple, optional) – Extra custom arguments for the progress callback function. You can pass anything you need to be available in the progress callback scope; for example, a Message object or a Client instance in order to edit the message with the updated progress status.

    Other Parameters:

            current (int) – The amount of bytes transmitted so far.

            total (int) – The total size of the file.

            *args (tuple, optional) – Extra custom arguments as defined in the progress_args parameter. You can either keep *args or add every single extra argument in your function signature.

    Returns:

        Message | None – On success, the sent photo message is returned, otherwise, in case the upload is deliberately stopped with stop_transmission(), None is returned.

    Example

    # Send photo by uploading from local file
    await app.send_photo("me", "photo.jpg")

    # Send photo by uploading from URL
    await app.send_photo("me", "https://example.com/example.jpg")

    # Add caption to a photo
    await app.send_photo("me", "photo.jpg", caption="Caption")

    # Send self-destructing photo
    await app.send_photo("me", "photo.jpg", ttl_seconds=10)

    # Send view-once photo
    await app.send_photo("me", "photo.jpg", view_once=True)


docs.kurigram.live
send_audio() - Kurigram
5 - 6 minutes

Toggle table of contents sidebar

Client.send_audio()¶

    Send audio files.

    For sending voice messages, use the send_voice() method instead.
    Usable by Users Bots

    Parameters:

            chat_id (int | str) – Unique identifier (int) or username (str) of the target chat. For your personal cloud (Saved Messages) you can simply use “me” or “self”. For a contact that exists in your Telegram address book you can use his phone number (str).

            audio (str | BinaryIO) – Audio file to send. Pass a file_id as string to send an audio file that exists on the Telegram servers, pass an HTTP URL as a string for Telegram to get an audio file from the Internet, pass a file path as string to upload a new audio file that exists on your local machine, or pass a binary file-like object with its attribute “.name” set for in-memory uploads.

            caption (str, optional) – Audio caption, 0-1024 characters.

            parse_mode (ParseMode, optional) – By default, texts are parsed using both Markdown and HTML styles. You can combine both syntaxes together.

            caption_entities (List of MessageEntity) – List of special entities that appear in the caption, which can be specified instead of parse_mode.

            duration (int, optional) – Duration of the audio in seconds.

            performer (str, optional) – Performer.

            title (str, optional) – Track name.

            thumb (str | BinaryIO, optional) – Thumbnail of the music file album cover. The thumbnail should be in JPEG format and less than 200 KB in size. A thumbnail’s width and height should not exceed 320 pixels. Thumbnails can’t be reused and can be only uploaded as a new file.

            file_name (str, optional) – File name of the audio sent. Defaults to file’s path basename.

            disable_notification (bool, optional) – Sends the message silently. Users will receive a notification with no sound.

            message_thread_id (int, optional) – Unique identifier for the target message thread (topic) of the forum. For forums only.

            direct_messages_topic_id (int, optional) – Unique identifier of the topic in a channel direct messages chat administered by the current user. For directs only only.

            effect_id (int, optional) – Unique identifier of the message effect. For private chats only.

            reply_parameters (ReplyParameters, optional) – Describes reply parameters for the message that is being sent.

            schedule_date (datetime, optional) – Date when the message will be automatically sent.

            protect_content (bool, optional) – Protects the contents of the sent message from forwarding and saving.

            business_connection_id (str, optional) – Unique identifier of the business connection on behalf of which the message will be sent.

            allow_paid_broadcast (bool, optional) – If True, you will be allowed to send up to 1000 messages per second. Ignoring broadcasting limits for a fee of 0.1 Telegram Stars per message. The relevant Stars will be withdrawn from the bot’s balance. For bots only.

            paid_message_star_count (int, optional) – The number of Telegram Stars the user agreed to pay to send the messages.

            suggested_post_parameters (SuggestedPostParameters, optional) – Information about the suggested post.

            reply_markup (InlineKeyboardMarkup | ReplyKeyboardMarkup | ReplyKeyboardRemove | ForceReply, optional) – Additional interface options. An object for an inline keyboard, custom reply keyboard, instructions to remove reply keyboard or to force a reply from the user.

            progress (Callable, optional) – Pass a callback function to view the file transmission progress. The function must take (current, total) as positional arguments (look at Other Parameters below for a detailed description) and will be called back each time a new file chunk has been successfully transmitted.

            progress_args (tuple, optional) – Extra custom arguments for the progress callback function. You can pass anything you need to be available in the progress callback scope; for example, a Message object or a Client instance in order to edit the message with the updated progress status.

    Other Parameters:

            current (int) – The amount of bytes transmitted so far.

            total (int) – The total size of the file.

            *args (tuple, optional) – Extra custom arguments as defined in the progress_args parameter. You can either keep *args or add every single extra argument in your function signature.

    Returns:

        Message | None – On success, the sent audio message is returned, otherwise, in case the upload is deliberately stopped with stop_transmission(), None is returned.

    Example

    # Send audio file by uploading from file
    await app.send_audio("me", "audio.mp3")

    # Add caption to the audio
    await app.send_audio("me", "audio.mp3", caption="audio caption")

    # Set audio metadata
    await app.send_audio(
        "me", "audio.mp3",
        title="Title", performer="Performer", duration=234)

    # Keep track of the progress while uploading
    async def progress(current, total):
        print(f"{current * 100 / total:.1f}%")

    await app.send_audio("me", "audio.mp3", progress=progress)


docs.kurigram.live
send_document() - Kurigram
5 - 6 minutes

Toggle table of contents sidebar

Client.send_document()¶

    Send generic files.
    Usable by Users Bots

    Parameters:

            chat_id (int | str) – Unique identifier (int) or username (str) of the target chat. For your personal cloud (Saved Messages) you can simply use “me” or “self”. For a contact that exists in your Telegram address book you can use his phone number (str).

            document (str | BinaryIO) – File to send. Pass a file_id as string to send a file that exists on the Telegram servers, pass an HTTP URL as a string for Telegram to get a file from the Internet, pass a file path as string to upload a new file that exists on your local machine, or pass a binary file-like object with its attribute “.name” set for in-memory uploads.

            thumb (str | BinaryIO, optional) – Thumbnail of the file sent. The thumbnail should be in JPEG format and less than 200 KB in size. A thumbnail’s width and height should not exceed 320 pixels. Thumbnails can’t be reused and can be only uploaded as a new file.

            caption (str, optional) – Document caption, 0-1024 characters.

            parse_mode (ParseMode, optional) – By default, texts are parsed using both Markdown and HTML styles. You can combine both syntaxes together.

            caption_entities (List of MessageEntity) – List of special entities that appear in the caption, which can be specified instead of parse_mode.

            file_name (str, optional) – File name of the document sent. Defaults to file’s path basename.

            force_document (bool, optional) – Pass True to force sending files as document. Useful for video files that need to be sent as document messages instead of video messages. Defaults to False.

            disable_notification (bool, optional) – Sends the message silently. Users will receive a notification with no sound.

            message_thread_id (int, optional) – Unique identifier for the target message thread (topic) of the forum. For forums only.

            direct_messages_topic_id (int, optional) – Unique identifier of the topic in a channel direct messages chat administered by the current user. For directs only only.

            effect_id (int, optional) – Unique identifier of the message effect. For private chats only.

            reply_parameters (ReplyParameters, optional) – Describes reply parameters for the message that is being sent.

            schedule_date (datetime, optional) – Date when the message will be automatically sent.

            protect_content (bool, optional) – Protects the contents of the sent message from forwarding and saving.

            business_connection_id (str, optional) – Unique identifier of the business connection on behalf of which the message will be sent.

            allow_paid_broadcast (bool, optional) – If True, you will be allowed to send up to 1000 messages per second. Ignoring broadcasting limits for a fee of 0.1 Telegram Stars per message. The relevant Stars will be withdrawn from the bot’s balance. For bots only.

            paid_message_star_count (int, optional) – The number of Telegram Stars the user agreed to pay to send the messages.

            suggested_post_parameters (SuggestedPostParameters, optional) – Information about the suggested post.

            reply_markup (InlineKeyboardMarkup | ReplyKeyboardMarkup | ReplyKeyboardRemove | ForceReply, optional) – Additional interface options. An object for an inline keyboard, custom reply keyboard, instructions to remove reply keyboard or to force a reply from the user.

            progress (Callable, optional) – Pass a callback function to view the file transmission progress. The function must take (current, total) as positional arguments (look at Other Parameters below for a detailed description) and will be called back each time a new file chunk has been successfully transmitted.

            progress_args (tuple, optional) – Extra custom arguments for the progress callback function. You can pass anything you need to be available in the progress callback scope; for example, a Message object or a Client instance in order to edit the message with the updated progress status.

    Other Parameters:

            current (int) – The amount of bytes transmitted so far.

            total (int) – The total size of the file.

            *args (tuple, optional) – Extra custom arguments as defined in the progress_args parameter. You can either keep *args or add every single extra argument in your function signature.

    Returns:

        Message | None – On success, the sent document message is returned, otherwise, in case the upload is deliberately stopped with stop_transmission(), None is returned.

    Example

    # Send document by uploading from local file
    await app.send_document("me", "document.zip")

    # Add caption to the document file
    await app.send_document("me", "document.zip", caption="document caption")

    # Keep track of the progress while uploading
    async def progress(current, total):
        print(f"{current * 100 / total:.1f}%")

    await app.send_document("me", "document.zip", progress=progress)


docs.kurigram.live
send_sticker() - Kurigram
4 - 5 minutes

Toggle table of contents sidebar

Client.send_sticker()¶

    Send static .webp or animated .tgs stickers.
    Usable by Users Bots

    Parameters:

            chat_id (int | str) – Unique identifier (int) or username (str) of the target chat. For your personal cloud (Saved Messages) you can simply use “me” or “self”. For a contact that exists in your Telegram address book you can use his phone number (str).

            sticker (str | BinaryIO) – Sticker to send. Pass a file_id as string to send a sticker that exists on the Telegram servers, pass an HTTP URL as a string for Telegram to get a .webp sticker file from the Internet, pass a file path as string to upload a new sticker that exists on your local machine, or pass a binary file-like object with its attribute “.name” set for in-memory uploads.

            emoji (str, optional) – Emoji associated with this sticker.

            caption (str, optional) – Sticker caption, 0-1024 characters.

            parse_mode (ParseMode, optional) – By default, texts are parsed using both Markdown and HTML styles. You can combine both syntaxes together.

            caption_entities (List of MessageEntity) – List of special entities that appear in the caption, which can be specified instead of parse_mode.

            disable_notification (bool, optional) – Sends the message silently. Users will receive a notification with no sound.

            message_thread_id (int, optional) – Unique identifier for the target message thread (topic) of the forum. For forums only.

            direct_messages_topic_id (int, optional) – Unique identifier of the topic in a channel direct messages chat administered by the current user. For directs only only.

            effect_id (int, optional) – Unique identifier of the message effect. For private chats only.

            reply_parameters (ReplyParameters, optional) – Describes reply parameters for the message that is being sent.

            schedule_date (datetime, optional) – Date when the message will be automatically sent.

            protect_content (bool, optional) – Protects the contents of the sent message from forwarding and saving.

            business_connection_id (str, optional) – Unique identifier of the business connection on behalf of which the message will be sent.

            allow_paid_broadcast (bool, optional) – If True, you will be allowed to send up to 1000 messages per second. Ignoring broadcasting limits for a fee of 0.1 Telegram Stars per message. The relevant Stars will be withdrawn from the bot’s balance. For bots only.

            paid_message_star_count (int, optional) – The number of Telegram Stars the user agreed to pay to send the messages.

            suggested_post_parameters (SuggestedPostParameters, optional) – Information about the suggested post.

            reply_markup (InlineKeyboardMarkup | ReplyKeyboardMarkup | ReplyKeyboardRemove | ForceReply, optional) – Additional interface options. An object for an inline keyboard, custom reply keyboard, instructions to remove reply keyboard or to force a reply from the user.

            progress (Callable, optional) – Pass a callback function to view the file transmission progress. The function must take (current, total) as positional arguments (look at Other Parameters below for a detailed description) and will be called back each time a new file chunk has been successfully transmitted.

            progress_args (tuple, optional) – Extra custom arguments for the progress callback function. You can pass anything you need to be available in the progress callback scope; for example, a Message object or a Client instance in order to edit the message with the updated progress status.

    Other Parameters:

            current (int) – The amount of bytes transmitted so far.

            total (int) – The total size of the file.

            *args (tuple, optional) – Extra custom arguments as defined in the progress_args parameter. You can either keep *args or add every single extra argument in your function signature.

    Returns:

        Message | None – On success, the sent sticker message is returned, otherwise, in case the upload is deliberately stopped with stop_transmission(), None is returned.

    Example

    # Send sticker by uploading from local file
    await app.send_sticker("me", "sticker.webp")

    # Send sticker using file_id
    await app.send_sticker("me", file_id)


docs.kurigram.live
send_video() - Kurigram
6 - 8 minutes

Toggle table of contents sidebar

Client.send_video()¶

    Send video files.

    Note

    Starting December 1, 2024 messages with video that are sent, copied or forwarded to groups and channels with a sufficiently large audience can be automatically scheduled by the server until the respective video is reencoded. Such messages will have scheduled property set and beware of using the correct message identifiers when using such Message objects.
    Usable by Users Bots

    Parameters:

            chat_id (int | str) – Unique identifier (int) or username (str) of the target chat. For your personal cloud (Saved Messages) you can simply use “me” or “self”. For a contact that exists in your Telegram address book you can use his phone number (str).

            video (str | BinaryIO) – Video to send. Pass a file_id as string to send a video that exists on the Telegram servers, pass an HTTP URL as a string for Telegram to get a video from the Internet, pass a file path as string to upload a new video that exists on your local machine, or pass a binary file-like object with its attribute “.name” set for in-memory uploads.

            caption (str, optional) – Video caption, 0-1024 characters.

            parse_mode (ParseMode, optional) – By default, texts are parsed using both Markdown and HTML styles. You can combine both syntaxes together.

            caption_entities (List of MessageEntity) – List of special entities that appear in the caption, which can be specified instead of parse_mode.

            has_spoiler (bool, optional) – Pass True if the video needs to be covered with a spoiler animation.

            ttl_seconds (int, optional) – Self-Destruct Timer. If you set a timer, the video will self-destruct in ttl_seconds seconds after it was viewed.

            view_once (bool, optional) – Self-Destruct Timer. If True, the photo will self-destruct after it was viewed.

            duration (int, optional) – Duration of sent video in seconds.

            width (int, optional) – Video width.

            height (int, optional) – Video height.

            video_start_timestamp (int, optional) – Video startpoint, in seconds.

            video_cover (str | BinaryIO, optional) – Video cover. Pass a file_id as string to attach a photo that exists on the Telegram servers, pass an HTTP URL as a string for Telegram to get a photo from the Internet, pass a file path as string to upload a new photo that exists on your local machine, or pass a binary file-like object with its attribute “.name” set for in-memory uploads.

            thumb (str | BinaryIO, optional) – Thumbnail of the video sent. The thumbnail should be in JPEG format and less than 200 KB in size. A thumbnail’s width and height should not exceed 320 pixels. Thumbnails can’t be reused and can be only uploaded as a new file.

            file_name (str, optional) – File name of the video sent. Defaults to file’s path basename.

            supports_streaming (bool, optional) – Pass True, if the uploaded video is suitable for streaming. Defaults to True.

            disable_notification (bool, optional) – Sends the message silently. Users will receive a notification with no sound.

            message_thread_id (int, optional) – Unique identifier for the target message thread (topic) of the forum. For forums only.

            direct_messages_topic_id (int, optional) – Unique identifier of the topic in a channel direct messages chat administered by the current user. For directs only only.

            effect_id (int, optional) – Unique identifier of the message effect. For private chats only.

            show_caption_above_media (bool, optional) – Pass True, if the caption must be shown above the message media.

            reply_parameters (ReplyParameters, optional) – Describes reply parameters for the message that is being sent.

            schedule_date (datetime, optional) – Date when the message will be automatically sent.

            protect_content (bool, optional) – Protects the contents of the sent message from forwarding and saving.

            no_sound (bool, optional) – Pass True, if the uploaded video is a video message with no sound. Doesn’t work for external links.

            business_connection_id (str, optional) – Unique identifier of the business connection on behalf of which the message will be sent.

            allow_paid_broadcast (bool, optional) – If True, you will be allowed to send up to 1000 messages per second. Ignoring broadcasting limits for a fee of 0.1 Telegram Stars per message. The relevant Stars will be withdrawn from the bot’s balance. For bots only.

            paid_message_star_count (int, optional) – The number of Telegram Stars the user agreed to pay to send the messages.

            suggested_post_parameters (SuggestedPostParameters, optional) – Information about the suggested post.

            reply_markup (InlineKeyboardMarkup | ReplyKeyboardMarkup | ReplyKeyboardRemove | ForceReply, optional) – Additional interface options. An object for an inline keyboard, custom reply keyboard, instructions to remove reply keyboard or to force a reply from the user.

            progress (Callable, optional) – Pass a callback function to view the file transmission progress. The function must take (current, total) as positional arguments (look at Other Parameters below for a detailed description) and will be called back each time a new file chunk has been successfully transmitted.

            progress_args (tuple, optional) – Extra custom arguments for the progress callback function. You can pass anything you need to be available in the progress callback scope; for example, a Message object or a Client instance in order to edit the message with the updated progress status.

    Other Parameters:

            current (int) – The amount of bytes transmitted so far.

            total (int) – The total size of the file.

            *args (tuple, optional) – Extra custom arguments as defined in the progress_args parameter. You can either keep *args or add every single extra argument in your function signature.

    Returns:

        Message | None – On success, the sent video message is returned, otherwise, in case the upload is deliberately stopped with stop_transmission(), None is returned.

    Example

    # Send video by uploading from local file
    await app.send_video("me", "video.mp4")

    # Add caption to the video
    await app.send_video("me", "video.mp4", caption="video caption")

    # Send self-destructing video
    await app.send_video("me", "video.mp4", ttl_seconds=10)

    # Send view-once video
    await app.send_video("me", "video.mp4", view_once=True)

    # Add video_cover to the video
    await app.send_video(channel_id, "video.mp4", video_cover="photo.jpg")

    # Keep track of the progress while uploading
    async def progress(current, total):
        print(f"{current * 100 / total:.1f}%")

    await app.send_video("me", "video.mp4", progress=progress)


docs.kurigram.live
send_animation() - Kurigram
5 - 7 minutes

Toggle table of contents sidebar

Client.send_animation()¶

    Send animation files (animation or H.264/MPEG-4 AVC video without sound).
    Usable by Users Bots

    Parameters:

            chat_id (int | str) – Unique identifier (int) or username (str) of the target chat. For your personal cloud (Saved Messages) you can simply use “me” or “self”. For a contact that exists in your Telegram address book you can use his phone number (str).

            animation (str | BinaryIO) – Animation to send. Pass a file_id as string to send an animation that exists on the Telegram servers, pass an HTTP URL as a string for Telegram to get an animation from the Internet, pass a file path as string to upload a new animation that exists on your local machine, or pass a binary file-like object with its attribute “.name” set for in-memory uploads.

            caption (str, optional) – Animation caption, 0-1024 characters.

            unsave (bool, optional) – By default, the server will save into your own collection any new animation you send. Pass True to automatically unsave the sent animation. Defaults to False.

            parse_mode (ParseMode, optional) – By default, texts are parsed using both Markdown and HTML styles. You can combine both syntaxes together.

            caption_entities (List of MessageEntity) – List of special entities that appear in the caption, which can be specified instead of parse_mode.

            has_spoiler (bool, optional) – Pass True if the animation needs to be covered with a spoiler animation.

            duration (int, optional) – Duration of sent animation in seconds.

            width (int, optional) – Animation width.

            height (int, optional) – Animation height.

            thumb (str | BinaryIO, optional) – Thumbnail of the animation file sent. The thumbnail should be in JPEG format and less than 200 KB in size. A thumbnail’s width and height should not exceed 320 pixels. Thumbnails can’t be reused and can be only uploaded as a new file.

            file_name (str, optional) – File name of the animation sent. Defaults to file’s path basename.

            disable_notification (bool, optional) – Sends the message silently. Users will receive a notification with no sound.

            message_thread_id (int, optional) – Unique identifier for the target message thread (topic) of the forum. For forums only.

            direct_messages_topic_id (int, optional) – Unique identifier of the topic in a channel direct messages chat administered by the current user. For directs only only.

            effect_id (int, optional) – Unique identifier of the message effect. For private chats only.

            show_caption_above_media (bool, optional) – Pass True, if the caption must be shown above the message media.

            reply_parameters (ReplyParameters, optional) – Describes reply parameters for the message that is being sent.

            schedule_date (datetime, optional) – Date when the message will be automatically sent.

            protect_content (bool, optional) – Protects the contents of the sent message from forwarding and saving.

            business_connection_id (str, optional) – Unique identifier of the business connection on behalf of which the message will be sent.

            allow_paid_broadcast (bool, optional) – If True, you will be allowed to send up to 1000 messages per second. Ignoring broadcasting limits for a fee of 0.1 Telegram Stars per message. The relevant Stars will be withdrawn from the bot’s balance. For bots only.

            paid_message_star_count (int, optional) – The number of Telegram Stars the user agreed to pay to send the messages.

            suggested_post_parameters (SuggestedPostParameters, optional) – Information about the suggested post.

            reply_markup (InlineKeyboardMarkup | ReplyKeyboardMarkup | ReplyKeyboardRemove | ForceReply, optional) – Additional interface options. An object for an inline keyboard, custom reply keyboard, instructions to remove reply keyboard or to force a reply from the user.

            progress (Callable, optional) – Pass a callback function to view the file transmission progress. The function must take (current, total) as positional arguments (look at Other Parameters below for a detailed description) and will be called back each time a new file chunk has been successfully transmitted.

            progress_args (tuple, optional) – Extra custom arguments for the progress callback function. You can pass anything you need to be available in the progress callback scope; for example, a Message object or a Client instance in order to edit the message with the updated progress status.

    Other Parameters:

            current (int) – The amount of bytes transmitted so far.

            total (int) – The total size of the file.

            *args (tuple, optional) – Extra custom arguments as defined in the progress_args parameter. You can either keep *args or add every single extra argument in your function signature.

    Returns:

        Message | None – On success, the sent animation message is returned, otherwise, in case the upload is deliberately stopped with stop_transmission(), None is returned.

    Example

    # Send animation by uploading from local file
    await app.send_animation("me", "animation.gif")

    # Add caption to the animation
    await app.send_animation("me", "animation.gif", caption="animation caption")

    # Unsave the animation once is sent
    await app.send_animation("me", "animation.gif", unsave=True)

    # Keep track of the progress while uploading
    async def progress(current, total):
        print(f"{current * 100 / total:.1f}%")

    await app.send_animation("me", "animation.gif", progress=progress)


docs.kurigram.live
send_voice() - Kurigram
5 - 6 minutes

Toggle table of contents sidebar

Client.send_voice()¶

    Send audio files.
    Usable by Users Bots

    Parameters:

            chat_id (int | str) – Unique identifier (int) or username (str) of the target chat. For your personal cloud (Saved Messages) you can simply use “me” or “self”. For a contact that exists in your Telegram address book you can use his phone number (str).

            voice (str | BinaryIO) – Audio file to send. Pass a file_id as string to send an audio that exists on the Telegram servers, pass an HTTP URL as a string for Telegram to get an audio from the Internet, pass a file path as string to upload a new audio that exists on your local machine, or pass a binary file-like object with its attribute “.name” set for in-memory uploads.

            caption (str, optional) – Voice message caption, 0-1024 characters.

            parse_mode (ParseMode, optional) – By default, texts are parsed using both Markdown and HTML styles. You can combine both syntaxes together.

            caption_entities (List of MessageEntity) – List of special entities that appear in the caption, which can be specified instead of parse_mode.

            duration (int, optional) – Duration of the voice message in seconds.

            disable_notification (bool, optional) – Sends the message silently. Users will receive a notification with no sound.

            message_thread_id (int, optional) – Unique identifier for the target message thread (topic) of the forum. For forums only.

            direct_messages_topic_id (int, optional) – Unique identifier of the topic in a channel direct messages chat administered by the current user. For directs only only.

            effect_id (int, optional) – Unique identifier of the message effect. For private chats only.

            reply_parameters (ReplyParameters, optional) – Describes reply parameters for the message that is being sent.

            schedule_date (datetime, optional) – Date when the message will be automatically sent.

            protect_content (bool, optional) – Protects the contents of the sent message from forwarding and saving.

            view_once (bool, optional) – Self-Destruct Timer. If True, the voice note will self-destruct after it was listened.

            business_connection_id (str, optional) – Unique identifier of the business connection on behalf of which the message will be sent.

            allow_paid_broadcast (bool, optional) – If True, you will be allowed to send up to 1000 messages per second. Ignoring broadcasting limits for a fee of 0.1 Telegram Stars per message. The relevant Stars will be withdrawn from the bot’s balance. For bots only.

            paid_message_star_count (int, optional) – The number of Telegram Stars the user agreed to pay to send the messages.

            suggested_post_parameters (SuggestedPostParameters, optional) – Information about the suggested post.

            reply_markup (InlineKeyboardMarkup | ReplyKeyboardMarkup | ReplyKeyboardRemove | ForceReply, optional) – Additional interface options. An object for an inline keyboard, custom reply keyboard, instructions to remove reply keyboard or to force a reply from the user.

            progress (Callable, optional) – Pass a callback function to view the file transmission progress. The function must take (current, total) as positional arguments (look at Other Parameters below for a detailed description) and will be called back each time a new file chunk has been successfully transmitted.

            progress_args (tuple, optional) – Extra custom arguments for the progress callback function. You can pass anything you need to be available in the progress callback scope; for example, a Message object or a Client instance in order to edit the message with the updated progress status.

    Other Parameters:

            current (int) – The amount of bytes transmitted so far.

            total (int) – The total size of the file.

            *args (tuple, optional) – Extra custom arguments as defined in the progress_args parameter. You can either keep *args or add every single extra argument in your function signature.

    Returns:

        Message | None – On success, the sent voice message is returned, otherwise, in case the upload is deliberately stopped with stop_transmission(), None is returned.

    Example

    # Send voice note by uploading from local file
    await app.send_voice("me", "voice.ogg")

    # Add caption to the voice note
    await app.send_voice("me", "voice.ogg", caption="voice caption")

    # Set voice note duration
    await app.send_voice("me", "voice.ogg", duration=20)

    # Send self-destructing voice note
    await app.send_voice("me", "voice.ogg", view_once=True)


docs.kurigram.live
send_video_note() - Kurigram
5 - 6 minutes

Toggle table of contents sidebar

Client.send_video_note()¶

    Send video messages.
    Usable by Users Bots

    Parameters:

            chat_id (int | str) – Unique identifier (int) or username (str) of the target chat. For your personal cloud (Saved Messages) you can simply use “me” or “self”. For a contact that exists in your Telegram address book you can use his phone number (str).

            video_note (str | BinaryIO) – Video note to send. Pass a file_id as string to send a video note that exists on the Telegram servers, pass a file path as string to upload a new video note that exists on your local machine, or pass a binary file-like object with its attribute “.name” set for in-memory uploads. Sending video notes by a URL is currently unsupported.

            Note

            When uploading from local file: if the file is larger than 10 MB, Telegram will upload it as a regular video instead of a video note.

            duration (int, optional) – Duration of sent video in seconds.

            length (int, optional) – Video width and height.

            thumb (str | BinaryIO, optional) – Thumbnail of the video sent. The thumbnail should be in JPEG format and less than 200 KB in size. A thumbnail’s width and height should not exceed 320 pixels. Thumbnails can’t be reused and can be only uploaded as a new file.

            disable_notification (bool, optional) – Sends the message silently. Users will receive a notification with no sound.

            message_thread_id (int, optional) – Unique identifier for the target message thread (topic) of the forum. For forums only.

            direct_messages_topic_id (int, optional) – Unique identifier of the topic in a channel direct messages chat administered by the current user. For directs only only.

            effect_id (int, optional) – Unique identifier of the message effect. For private chats only.

            reply_parameters (ReplyParameters, optional) – Describes reply parameters for the message that is being sent.

            schedule_date (datetime, optional) – Date when the message will be automatically sent.

            protect_content (bool, optional) – Protects the contents of the sent message from forwarding and saving.

            view_once (bool, optional) – Self-Destruct Timer. If True, the video note will self-destruct after it was viewed.

            business_connection_id (str, optional) – Unique identifier of the business connection on behalf of which the message will be sent.

            allow_paid_broadcast (bool, optional) – If True, you will be allowed to send up to 1000 messages per second. Ignoring broadcasting limits for a fee of 0.1 Telegram Stars per message. The relevant Stars will be withdrawn from the bot’s balance. For bots only.

            paid_message_star_count (int, optional) – The number of Telegram Stars the user agreed to pay to send the messages.

            suggested_post_parameters (SuggestedPostParameters, optional) – Information about the suggested post.

            reply_markup (InlineKeyboardMarkup | ReplyKeyboardMarkup | ReplyKeyboardRemove | ForceReply, optional) – Additional interface options. An object for an inline keyboard, custom reply keyboard, instructions to remove reply keyboard or to force a reply from the user.

            progress (Callable, optional) – Pass a callback function to view the file transmission progress. The function must take (current, total) as positional arguments (look at Other Parameters below for a detailed description) and will be called back each time a new file chunk has been successfully transmitted.

            progress_args (tuple, optional) – Extra custom arguments for the progress callback function. You can pass anything you need to be available in the progress callback scope; for example, a Message object or a Client instance in order to edit the message with the updated progress status.

    Other Parameters:

            current (int) – The amount of bytes transmitted so far.

            total (int) – The total size of the file.

            *args (tuple, optional) – Extra custom arguments as defined in the progress_args parameter. You can either keep *args or add every single extra argument in your function signature.

    Returns:

        Message | None – On success, the sent video note message is returned, otherwise, in case the upload is deliberately stopped with stop_transmission(), None is returned.

    Example

    # Send video note by uploading from local file
    await app.send_video_note("me", "video_note.mp4")

    # Set video note length
    await app.send_video_note("me", "video_note.mp4", length=25)

    # Send self-destructing video note
    await app.send_video_note("me", "video_note.mp4", view_once=True)


docs.kurigram.live
send_media_group() - Kurigram
3 minutes

Toggle table of contents sidebar

Client.send_media_group()¶

    Send a group of photos or videos as an album.
    Usable by Users Bots

    Parameters:

            chat_id (int | str) – Unique identifier (int) or username (str) of the target chat. For your personal cloud (Saved Messages) you can simply use “me” or “self”. For a contact that exists in your Telegram address book you can use his phone number (str).

            media (List of InputMediaPhoto, InputMediaVideo, InputMediaAudio and InputMediaDocument) – A list describing photos and videos to be sent, must include 2–10 items.

            disable_notification (bool, optional) – Sends the message silently. Users will receive a notification with no sound.

            message_thread_id (int, optional) – Unique identifier for the target message thread (topic) of the forum. For forums only.

            direct_messages_topic_id (int, optional) – Unique identifier of the topic in a channel direct messages chat administered by the current user. For directs only only.

            effect_id (int, optional) – Unique identifier of the message effect. For private chats only.

            reply_parameters (ReplyParameters, optional) – Describes reply parameters for the message that is being sent.

            schedule_date (datetime, optional) – Date when the message will be automatically sent.

            protect_content (bool, optional) – Protects the contents of the sent message from forwarding and saving.

            show_caption_above_media (bool, optional) – Pass True, if the caption must be shown above the message media.

            business_connection_id (str, optional) – Unique identifier of the business connection on behalf of which the message will be sent.

            allow_paid_broadcast (bool, optional) – If True, you will be allowed to send up to 1000 messages per second. Ignoring broadcasting limits for a fee of 0.1 Telegram Stars per message. The relevant Stars will be withdrawn from the bot’s balance. For bots only.

            paid_message_star_count (int, optional) – The number of Telegram Stars the user agreed to pay to send the messages.

    Returns:

        List of Message – On success, a list of the sent messages is returned.

    Example

    from pyrogram.types import InputMediaPhoto, InputMediaVideo

    await app.send_media_group(
        "me",
        [
            InputMediaPhoto("photo1.jpg"),
            InputMediaPhoto("photo2.jpg", caption="photo caption"),
            InputMediaVideo("video.mp4", caption="video caption")
        ]
    )


docs.kurigram.live
send_contact() - Kurigram
3 minutes

Toggle table of contents sidebar

Client.send_contact()¶

    Send phone contacts.
    Usable by Users Bots

    Parameters:

            chat_id (int | str) – Unique identifier (int) or username (str) of the target chat. For your personal cloud (Saved Messages) you can simply use “me” or “self”. For a contact that exists in your Telegram address book you can use his phone number (str).

            phone_number (str) – Contact’s phone number.

            first_name (str) – Contact’s first name.

            last_name (str, optional) – Contact’s last name.

            vcard (str, optional) – Additional data about the contact in the form of a vCard, 0-2048 bytes

            disable_notification (bool, optional) – Sends the message silently. Users will receive a notification with no sound.

            message_thread_id (int, optional) – Unique identifier for the target message thread (topic) of the forum. For forums only.

            direct_messages_topic_id (int, optional) – Unique identifier of the topic in a channel direct messages chat administered by the current user. For directs only only.

            effect_id (int, optional) – Unique identifier of the message effect. For private chats only.

            reply_parameters (ReplyParameters, optional) – Describes reply parameters for the message that is being sent.

            suggested_post_parameters (SuggestedPostParameters, optional) – Information about the suggested post.

            schedule_date (datetime, optional) – Date when the message will be automatically sent.

            protect_content (bool, optional) – Protects the contents of the sent message from forwarding and saving.

            business_connection_id (str, optional) – Unique identifier of the business connection on behalf of which the message will be sent.

            allow_paid_broadcast (bool, optional) – If True, you will be allowed to send up to 1000 messages per second. Ignoring broadcasting limits for a fee of 0.1 Telegram Stars per message. The relevant Stars will be withdrawn from the bot’s balance. For bots only.

            paid_message_star_count (int, optional) – The number of Telegram Stars the user agreed to pay to send the messages.

            reply_markup (InlineKeyboardMarkup | ReplyKeyboardMarkup | ReplyKeyboardRemove | ForceReply, optional) – Additional interface options. An object for an inline keyboard, custom reply keyboard, instructions to remove reply keyboard or to force a reply from the user.

    Returns:

        Message – On success, the sent contact message is returned.

    Example

    await app.send_contact("me", "+1-123-456-7890", "Name")

