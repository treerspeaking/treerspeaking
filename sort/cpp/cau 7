static void sortSegment(T* start, T* end, int segment_idx, int cur_segment_total) {
    // TODO
    int size = end - start;
    for (int curr = segment_idx + cur_segment_total; curr < size; curr += cur_segment_total) {
        int tmp = start[curr];
        int i;
        for (i = curr - cur_segment_total; i >= 0 && start[i] > tmp;
            i -= cur_segment_total) {
                start[i + cur_segment_total] = start[i];
            }
        start[i + cur_segment_total] = tmp;
    }
}

static void ShellSort(T* start, T* end, int* num_segment_list, int num_phases) {
    // TODO
    // Note: You must print out the array after sorting segments to check whether your algorithm is true.
    for (int phase = num_phases - 1; phase >= 0; phase--) {
        int step = num_segment_list[phase];
        for (int segment = 0; segment < step; segment++) {
            sortSegment(start, end, segment, step);
        }
        cout << step << " segments: ";
        printArray(start, end);
    }
}